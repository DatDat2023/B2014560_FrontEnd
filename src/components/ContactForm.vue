import React, { useState, useEffect } from 'react';

const ContactForm = ({ contact }) => {
  const [mode, setMode] = useState('add');
  
  useEffect(() => {
    if (contact && contact.id) {
      setMode('edit');
    }
  }, [contact]);

  const handleDelete = () => {
    // Xử lý logic xóa liên hệ
  };

  return (
    <div>
      <form>
        {/* Các trường dữ liệu của liên hệ */}
      </form>
      {mode === 'edit' && (
        <button onClick={handleDelete}>Xóa liên hệ</button>
      )}
    </div>
  );
};

export default ContactForm;
